# $NetBSD$
#

DISTNAME=		cclive-0.7.0b4
CATEGORIES=		net multimedia www
MASTER_SITES=		http://cclive.googlecode.com/files/
EXTRACT_SUFX=		.tar.bz2

MAINTAINER= 		ryo_on@yk.rim.or.jp
HOMEPAGE=		http://code.google.com/p/cclive/
COMMENT=		Command line video extraction tool for user-uploaded video hosts
LICENSE=		gnu-gpl-v3

PKG_DESTDIR_SUPPORT=	user-destdir

USE_LANGUAGES=		c++ c
USE_CMAKE=		yes
USE_TOOLS+=		pkg-config gmake

INSTALLATION_DIRS=	bin ${PKGMANDIR}/man1

CMAKE_ARGS+=		-DCMAKE_BUILD_TYPE=debug

#do-install:
#	${INSTALL_PROGRAM} ${WRKSRC}/src/cclive ${DESTDIR}${PREFIX}/bin
#	${INSTALL_MAN} ${WRKSRC}/cclive.1 ${DESTDIR}${PREFIX}/${PKGMANDIR}/man1

.include "../../wip/quvi/buildlink3.mk"
.include "../../www/curl/buildlink3.mk"
.include "../../devel/pcre++/buildlink3.mk"
.include "../../devel/boost-libs/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
