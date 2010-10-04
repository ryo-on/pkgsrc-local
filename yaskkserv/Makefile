# $NetBSD$
#

DISTNAME=	yaskkserv-0.4.0
CATEGORIES=	inputmethod japanese
MASTER_SITES=	http://umiushi.org/~wac/yaskkserv/
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://umiushi.org/~wac/yaskkserv/
COMMENT=	The small and fast SKK dictionary server intended for embedded use
LICENSE=	gnu-gpl-v2

PKG_DESTDIR_SUPPORT=	user-destdir

REPLACE_PERL=	configure

SUBST_CLASSES+=			proot
SUBST_STAGE.proot=		pre-configure
SUBST_MESSAGE.proot=		change ./ to WRKSRC
SUBST_FILES.proot=		configure
SUBST_SED.proot=		-e 's,Makefile.config,${WRKSRC}/Makefile.config,g'

SUBST_CLASSES+=			fix-paths
SUBST_STAGE.fix-paths=		pre-build
SUBST_MESSAGE.fix-paths=	PROJECTROOT to WRKSRC
SUBST_FILES.fix-paths=		Makefile.config
SUBST_SED.fix-paths=		-e 's,/usr/local,${DESTDIR}${PREFIX},g'
SUBST_SED.fix-paths+=		-e 's,^export PROJECT_ROOT.*,export PROJECT_ROOT = ${WRKSRC},g'


DEPENDS=	p5-Getopt-Long>=2.38:../../devel/p5-Getopt-Long
DEPENDS+=	p5-File-Temp>=0.22:../../devel/p5-File-Temp

USE_TOOLS+=	gmake perl:build
#HAS_CONFIGURE=	yes
USE_LANGUAGES=	c++

do-configure:
	${WRKSRC}/configure

.include "../../mk/bsd.pkg.mk"
