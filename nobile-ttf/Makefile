# $NetBSD$
#

DISTNAME=	Nobile
PKGNAME=	nobile-1
CATEGORIES=	fonts
MASTER_SITES=	http://ryo-on.users.sourceforge.net/distrib/fonts/
EXTRACT_SUFX=	.zip

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://www.fontsquirrel.com/fonts/Nobile
COMMENT=	Nobile is sans-serif font family
LICENSE=	open-font-license

PKG_DESTDIR_SUPPORT=	user-destdir

USE_X11BASE=	yes
NO_CONFIGURE=	yes
NO_BUILD=	yes

INSTALLATION_DIRS=	lib/X11/fonts/TTF

FONTDIR=	${PREFIX}/lib/X11/fonts/TTF
FONTS_DIRS.ttf=	${FONTDIR}

INSTALL_FONTS=	nobile.ttf \
		nobile_italic.ttf \
		nobile_bold.ttf \
		nobile_bold_italic.ttf

USE_LANGUAGES=	# none

WRKSRC=	${WRKDIR}

do-install:
.for fontfile in ${INSTALL_FONTS}
	${INSTALL_DATA} ${WRKSRC}/${fontfile} ${DESTDIR}${FONTDIR}
.endfor

.include "../../mk/bsd.pkg.mk"
