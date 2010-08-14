# $NetBSD$
#

DISTNAME=	juvelo-1.0
CATEGORIES=	fonts
MASTER_SITES=	http://crudfactory.com/cf3/fonts/
EXTRACT_SUFX=	.zip

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://crudfactory.com/cf3/juvelo.xhtml
COMMENT=	Juvelo font
LICENSE=	public-domain

PKG_DESTDIR_SUPPORT=	user-destdir

WRKSRC=		${WRKDIR}
USE_LANGUAGES=	# none
USE_X11BASE=	YES
NO_BUILD=	YES

FONTDIR=	${PREFIX}/lib/X11/fonts/TTF
FONTS_DIRS.ttf=	${FONTDIR}

INSTALLATION_DIRS=	lib/X11/fonts/TTF \
			${DOCSDIR}

INSTALL_FONTS=	Juvelo.otf

do-install:
.for filename in ${INSTALL_FONTS}
	${INSTALL_DATA} ${WRKSRC}/${filename} ${DESTDIR}${FONTDIR}
.endfor

.include "../../mk/bsd.pkg.mk"
